parse���ڴ�һ���ַ����н�����json����,��

var str = '{"name":"huangxiaojian","age":"23"}'

�����

JSON.parse(str)



Object

age: "23"
name: "huangxiaojian"
__proto__: Object



ע�⣺������д��{}�⣬ÿ����������������˫���ţ�������׳��쳣��



stringify()���ڴ�һ������������ַ�������


var
 a = {a:1,b:2}

�����

JSON.stringify(a)


"{"a":1,"b":2}"



//���鰴�ն�������
var compare = function (prop) {
    return function (obj1, obj2) {
        var val1 = obj1[prop];
        var val2 = obj2[prop];
        if (val1 < val2) {
            return -1;
        } else if (val1 > val2) {
            return 1;
        } else {
            return 0;
        }            
    } 
}
  datajs.sort(compare('agent_id'));