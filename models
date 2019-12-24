const N = 20;
const cellSize = 20;
const deadColor = "#000";
const liveColor = "#f1c40f"

let state = [];

for(let i = 0; i<N; i++){
state.push([]);
for(let j =0; j<N; j++){
state[i][j] = 0;
}
}

function stateTransition() {
let newState = [];
for(let i = 0; i<N; i++){
newState.push([]);
for(let j =0; j<N; j++){
newState[i][j] = 0;
}
}
for(let i = 0; i<N; i++){
for(let j = 0; j < N; j++){
let count = counter(i, j);

if(state[i][j] == 1){
if(count == 2 || count == 3) {
newState[i][j] = 1;
}
else{
newState[i][j] = 0;
}
}
if(state[i][j] == 0){
if(count == 3) {
newState[i][j] = 1;
}else{
newState[i][j] = 0
}
}


}
}

console.log(newState)
state = newState;
}

function isLive(i, j){
if(i < 0 || j < 0){
return 0;
}
if(i >= N || j >= N){
return 0;
}
return state[i][j];
}
function counter(i, j){
let k = 0;
if(isLive(i - 1, j - 1) == 1) {
k++;
}
if(isLive(i - 1, j) == 1) {
k++;
}
if(isLive(i - 1, j + 1) == 1) {
k++;
}
if(isLive(i, j - 1) == 1) {
k++;
}
if(isLive(i, j + 1) == 1) {
k++;
}
if(isLive(i + 1, j - 1) == 1) {
k++;
}
if(isLive(i + 1, j) == 1) {
k++;
}
if(isLive(i + 1, j + 1) == 1) {
k++;
}
return k;
}

function startLife(){

}
function gameStep() {
stateTransition();
coloring();

setTimeout(gameStep, 100);
}
