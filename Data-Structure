function total = femaleldlchdrisk(d) %struc array

%for patient's data find age within range
% p = patient , d = data

zeros(1,numel(d))
for p= 1:numel(d)

if d(p).age <= 34
    pts = -9;
elseif d(p).age >= 30 && d(p).age <= 34
    pts = -4;
elseif d(p).age >= 35 && d(p).age <= 39
    pts = 0;
elseif d(p).age >= 40 && d(p).age <= 44
    pts = 3;
elseif d(p).age >= 45 && d(p).age <= 49
    pts = 6;
elseif d(p).age >= 55 && d(p).age <= 59
    pts = 7;
elseif d(p).age >= 60 && d(p).age <= 74 || d(p).age > 74
    pts = 8;
end

if d(p).ldl < 100
    pts = -2;
elseif d(p).ldl < 190
    pts = 0;
elseif d(p).ldl >= 190
    pts = 2;
end
% for patient's hdl find within range
if d(p).hdl < 35
    pts = 5;
elseif d(p).hdl >= 35 &&  d(p).hdl <= 44
    pts = 2;
elseif d(p).hdl >= 45 &&  d(p).hdl <= 49
    pts = 1;
elseif d(p).hdl >= 50 &&  d(p).hdl <= 59
    pts = 0;
elseif d(p).hdl >= 60
    pts = -2;
end
% for range within bp
if d(p).systolic < 120 && d(p).diastolic < 80
    pts = -3;
elseif d(p).systolic >= 120 && d(p).systolic <= 139 && d(p).diastolic >= 80 && d(p).diastolic <= 84
    pts = 0;
elseif d(p).systolic >= 140 && d(p).systolic <= 159 && d(p).diastolic >= 85 && d(p).diastolic <= 89
    pts = 2;
elseif d(p).systolic >= 160 && d(p).diastolic >= 100
    pts = 3;
end

% if patient is a diabetic then true
if d(p).hasdiabetes == true
    pts = 4;
else
    pts = 0;
end

if d(p).issmoker == true
    pts = 2;
else
    pts = 0;
end

total = age + ldl + hdl + systolic + diastolic + hasdiabetes +issmoker;
end
