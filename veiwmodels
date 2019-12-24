
function tableClickHandler(ev) {
console.log('', ev.srcElement.id);
let id = parseInt(ev.srcElement.id);
let j = parseInt(id % N);
let i = parseInt(id / N);
if(state[i][j] == 1) state[i][j] = 0;
else state[i][j] = 1;
coloring();
}

function createUniverse() {
var body = document.getElementById('container');
var tbl = document.createElement('table');
tbl.style.width = cellSize*N + 'px';
tbl.style.height = cellSize*N + 'px';
tbl.className = "universeTable";
tbl.setAttribute('border', '1');
var tbdy = document.createElement('tbody');
for (var i = 0; i < N; i++) {
var tr = document.createElement('tr');
for (var j = 0; j < N; j++) {
var td = document.createElement('td');
td.id = `${i*N + j}`;
td.onclick = tableClickHandler;
tr.appendChild(td)
}
tbdy.appendChild(tr);
}
tbl.appendChild(tbdy);
body.appendChild(tbl)
coloring();
}
function coloring(){
for(let i = 0; i< N; i++){
for(let j = 0; j < N; j++){
let cell =document.getElementById(`${i*N+j}`);
if(state[i][j] == 0){
cell.style.backgroundColor = deadColor;
}
else{
cell.style.backgroundColor = liveColor;
}
}
}

}
