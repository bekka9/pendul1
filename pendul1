function [timeline, coords] = pendul1(rod1, theta1_0, timespan)
    l1 = rod1(1);
    m1 = rod1(2);
    g = 9.81; % ускорение свободного падения
    y0 = [theta1_0, 0]; % начальные условия
    time_step = 0.01;

    timeline = timespan(1):time_step:timespan(2);
    [t, y] = ode45(
      @(time,y) pendul1_ode(timeline,y,m1,l1,g), timeline, y0
    ); % решение системы ОДУ

    #смещение в декартовых координатах
    x1 = l1 * sin(y(:, 1));
    y1 = -l1 * cos(y(:, 1));

    #концы звеньев
    coords = [x1, y1];
end

function dydt = pendul1_ode(t,y,m1,l1,g)
    dydt = zeros(2,1);
    dydt(1) = y(2);
    dydt(2) = (-g*(2*m1)*sin(y(1)))/(l1*(2*m1));
end



