/**********������*******************/
/
/test����С�����м�㣬��arduino����ͨ�ţ�������������readme

roslaunch test arduino.launch


//���ֿ��Ʒ�ʽ�������Ƿ���x,y���ٶȣ�z�Ľ���
--------opencv

//������usb_cam,��������ͷ

roslaunch usb_cam usb_cam-test.launch

//����opencv���������

roslaunch opencvfinally 

---------����

teleop_twist_keyboard teleop_twist_keyboard.py


�����õ�С����************/

-------��鴮��
ls /dev/tty*


------��������ĳ����
catkin_make -DCATKIN_WHITELIST_PACKAGES="test"


-------�������
rqt_graph //��黰��֮��Ĺ�ϵ
rostopic list 
//��ʾ���л���
rostopic info XXXX //��ʾ��������֮�䶩���Լ�����


---------�ٶ����
rostopic pub /cmd_vel geometry_msgsros/Twist -r 1 -- '[2.0, 0.0, 0.0]' '[0.0, 0.0, 1.8]'

//�����ٶ�
rostopic echo /odom  ��

rosrun rqt_plot rqt_plot
ͼ�λ���ʾ��
/odom/pose/pose/orientation



