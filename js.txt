const tests = [];  

function addTest() {  
    const testNameInput = document.getElementById('test-name');  
    const testName = testNameInput.value.trim();  

    if (testName) {  
        tests.push(testName);  
        testNameInput.value = '';  
        renderTestList();  
    } else {  
        alert("يرجى إدخال اسم التحليل");  
    }  
}  

function renderTestList() {  
    const testList = document.getElementById('test-list');  
    testList.innerHTML = '';  

    tests.forEach((test, index) => {  
        const li = document.createElement('li');  
        li.textContent = `${index + 1}. ${test}`;  
        testList.appendChild(li);  
    });  
}