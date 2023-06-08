#параметры
m1 = 1;
l1 = 1;
rod1 = [l1 m1];

#отклонение
theta1_0 = pi/4;

timespan = [0, 10];

#моделирование движения маятника
[t, coords] = pendul1(rod1, theta1_0, timespan);

#анимация движения маятника
figure;
hold on;

pend1 = line('XData', [0 coords(1,1)], 'YData', [0 coords(1, 2)], 'LineWidth', 1);
ball_1_traect = line('XData', coords(1,1), 'YData', coords(1,2), 'Marker', 'o', 'MarkerFaceColor', 'b','MarkerSize', 4);
ball_1_traectline = line('XData', coords(:,1), 'YData', coords(:,2), 'LineWidth', 0.01, "color", "g");

axis([-2 2 -4 0]);

for i = 2:length(t)
    set(pend1, 'XData', [0 coords(i, 1)], 'YData', [0 coords(i, 2)]);
    set(ball_1_traect, 'XData', coords(i, 1), 'YData',coords(i, 2));
    set(ball_1_traectline, 'XData', coords(1:i, 1), 'YData',coords(1:i, 2));

    pause(0.01);
    drawnow;
    hold off;


end
