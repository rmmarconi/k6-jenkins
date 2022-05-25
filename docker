import http from 'k6/http';

export const options = {
  hosts: { 'rafaelmarconi.com.br': '66.70.177.16' },
  stages: [
    { duration: '1m', target: 10 },
    { duration: '1m', target: 20 },
    { duration: '1m', target: 10 },
  ],
  thresholds: { 
    http_req_duration: [
      { 
        threshold: 'avg<100', 
        threshold: 'p(95)<1500',
        abortOnFail: true,
      },
    ],
},
  noConnectionReuse: true,
  userAgent: 'MyK6UserAgentString/1.0',
};

export default function () {
  http.get('https://rafaelmarconi.com.br/');
}