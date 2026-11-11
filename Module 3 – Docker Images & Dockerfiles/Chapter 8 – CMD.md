
## Chapter 8 – CMD

Defines the default command when a container starts.

Example: `CMD ["python","app.py"]`

Only one CMD should exist.

If you write: 

```
CMD ["echo","First"]

CMD ["echo","Second"]
```

Only the last one runs.

Output: `Second`
